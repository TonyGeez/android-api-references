# AnimationDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationDrawable

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/AnimationDrawable "View this page in Java") 
| --- | --- |

```
open class AnimationDrawable : DrawableContainer, Animatable, Runnable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |||
| | ↳ | [android.graphics.drawable.DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer) ||
| | | ↳ | [android.graphics.drawable.AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#) |
| --- | --- | --- | --- |

An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background.

The simplest way to create a frame-by-frame animation is to define the animation in an XML file, placed in the res/drawable/ folder, and set it as the background to a View object. Then, call [start()](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#start())to run the animation.

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
| [`android:drawable`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#attr_AnimationDrawable) | Reference to a drawable resource to use for the frame. |
| [`android:duration`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#attr_AnimationDrawable) | Amount of time (in milliseconds) to display this frame. |
| [`android:oneshot`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#attr_AnimationDrawable) | If true, the animation will only run a single time and then stop. |
| --- | --- |
| [`android:variablePadding`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#attr_AnimationDrawable) | If true, allows the drawable's padding to change based on the current state that is selected. |
| [`android:visible`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#attr_AnimationDrawable) | Provides initial visibility state of the drawable; the default value is false. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#AnimationDrawable())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFrame](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#addFrame(android.graphics.drawable.Drawable,%20kotlin.Int))`(`frame:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a frame to the animation |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#getDuration(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)! | [getFrame](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#getFrame(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberOfFrames](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#getNumberOfFrames())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOneShot](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#isOneShot())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#isRunning())`()` Indicates whether the animation is currently running or not. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [mutate](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#mutate())`()` Make this drawable mutable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#run())`()` This method exists for implementation purpose only and should not be called directly. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOneShot](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#setOneShot(kotlin.Boolean))`(`oneShot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the animation should play once or repeat. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#setVisible(kotlin.Boolean,%20kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this AnimationDrawable is visible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#start())`()` Starts the animation from the first frame, looping if necessary. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#stop())`()` Stops the animation at the current frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#setConstantState(android.graphics.drawable.DrawableContainer.DrawableContainerState))`(`state:` ` [DrawableContainer.DrawableContainerState](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer.DrawableContainerState)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#applyTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#canApplyTheme())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getAlpha())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getChangingConfigurations())`()` <br /> Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | [getConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getConstantState())`()` <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [getCurrent](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getCurrent())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getHotspotBounds(android.graphics.Rect))`(`outRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getIntrinsicHeight())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getIntrinsicWidth())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getMinimumHeight())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getMinimumWidth())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOpacity())`()` <br /> | | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getOpticalInsets](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOpticalInsets())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getPadding(android.graphics.Rect))`(`padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#hasFocusStateSpecified())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#invalidateDrawable(android.graphics.drawable.Drawable))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`)` <br /> Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#isAutoMirrored())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#isStateful())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#jumpToCurrentState())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onBoundsChange(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onLayoutDirectionChanged(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onLevelChange(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onStateChange(kotlin.IntArray))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`, `what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call [android.os.Handler#postAtTime(Runnable, Object, long)](https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long))with the parameters (what, who, when) to perform the scheduling. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [selectDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#selectDrawable(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the currently displayed drawable by index. If an invalid index is specified, the current drawable will be set to`null`and the index will be set to`-1`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setAlpha(kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setAutoMirrored(kotlin.Boolean))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setColorFilter(android.graphics.ColorFilter))`(`colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setDither(kotlin.Boolean))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterFadeDuration](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setEnterFadeDuration(kotlin.Int))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is entering the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitFadeDuration](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setExitFadeDuration(kotlin.Int))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is leaving the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setHotspot(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`, `what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)). An implementation can generally simply call [android.os.Handler#removeCallbacks(Runnable, Object)](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any))with the parameters (what, who) to unschedule the drawable. <br /> | ||
| From class [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter())`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds())`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromPath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds())`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | [getCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback())`()` <br /> Return the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation attached to this Drawable. <br /> | | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | [getColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getColorFilter())`()` <br /> Returns the current color filter, or`null`if none set. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getDirtyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds())`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection())`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())`()` <br /> Retrieve the current level. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState())`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_selected](https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion())`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())`()` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected())`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback))`(`cb:` ` [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?`)` <br /> Bind a [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))which constructs a [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#). **Note:** Setting a color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_pressed](https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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
Provides initial visibility state of the drawable; the default value is false. See [android.graphics.drawable.Drawable#setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean)).

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
| `frame` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable):The frame to add This value cannot be`null`. |
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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)! | The Drawable at the specified frame index |

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
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#):Resources used to resolve attribute values This value cannot be`null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#):XML parser from which to inflate this Drawable This value cannot be`null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#):Base set of attribute values This value cannot be`null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?:Theme to apply, may be null |

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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | This value cannot be`null`. |

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun run(): Unit
```

This method exists for implementation purpose only and should not be called directly. Invoke [start()](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#start())instead. 
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

When the drawable becomes invisible, it will pause its animation. A subsequent change to visible with`restart`set to true will restart the animation from the first frame. If`restart`is false, the drawable will resume from the most recent frame. If the drawable has already reached the last frame, it will then loop back to the first frame, unless it's a one shot drawable (set through [setOneShot(boolean)](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#setOneShot(kotlin.Boolean))), in which case, it will stay on the last frame.

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

**Note:** Do not call this in the android.app.Activity#onCreate method of your activity, because the [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#) is not yet fully attached to the window. If you want to play the animation immediately without requiring interaction, then you might want to call it from the [android.app.Activity#onWindowFocusChanged](https://developer.android.com/reference/kotlin/android/app/Activity.html#onWindowFocusChanged(kotlin.Boolean))method in your activity, which will get called when Android brings your window into focus. 
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
| `what` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#):The runnable that you no longer want called. This value cannot be`null`. |

## Protected methods

### setConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setConstantState(state: DrawableContainer.DrawableContainerState): Unit
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [DrawableContainer.DrawableContainerState](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer.DrawableContainerState):This value cannot be`null`. |
