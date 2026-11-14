# AnimatedImageDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatedImageDrawable

Kotlin | [Java](../android/graphics/drawable/AnimatedImageDrawable.md) 
| --- | --- |

```
open class AnimatedImageDrawable : Drawable, Animatable2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](../android/graphics/drawable/Drawable.md) ||
| | ↳ | [android.graphics.drawable.AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md) |

[Drawable](../android/graphics/drawable/Drawable.md) for drawing animated images (like GIF).

The framework handles decoding subsequent frames in another thread and updating when necessary. The drawable will only animate while it is being displayed.

Created by android.graphics.ImageDecoder#decodeDrawable. A user needs to call [start](../android/graphics/drawable/AnimatedImageDrawable.md)) to start the animation.

It can also be defined in XML using the `<animated-image>` element.

## Summary

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [`android:autoMirrored`](../android/graphics/drawable/AnimatedImageDrawable.md) | Indicates if the drawable needs to be mirrored when its layout direction is RTL (right-to-left). |
| [`android:autoStart`](../android/graphics/drawable/AnimatedImageDrawable.md) | When true, automatically start animating. |
| [`android:repeatCount`](../android/graphics/drawable/AnimatedImageDrawable.md) | Replace the loop count in the encoded data. |
| --- | --- |
| [`android:src`](../android/graphics/drawable/AnimatedImageDrawable.md) | Identifier of the image file. |

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPEAT_INFINITE](../android/graphics/drawable/AnimatedImageDrawable.md) Pass this to [setRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md)) to repeat infinitely. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Create an empty AnimatedImageDrawable. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAnimationCallbacks](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/drawable/AnimatedImageDrawable.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| --- | --- |
| open [ColorFilter](../android/graphics/ColorFilter.md)? | [getColorFilter](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Returns the current color filter, or `null` if none set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Return the opacity/transparency of this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Retrieve the number of times the animation will repeat. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/graphics/drawable/AnimatedImageDrawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](../android/graphics/drawable/AnimatedImageDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Return whether the animation is currently running. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](../android/graphics/drawable/AnimatedImageDrawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAnimationCallback](../android/graphics/drawable/AnimatedImageDrawable.md))`(`callback:` ` [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md)`)` Adds a callback to listen to the animation events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](../android/graphics/drawable/AnimatedImageDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify an alpha value for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](../android/graphics/drawable/AnimatedImageDrawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](../android/graphics/drawable/AnimatedImageDrawable.md))`(`colorFilter:` ` [ColorFilter](../android/graphics/ColorFilter.md)?`)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](../android/graphics/drawable/AnimatedImageDrawable.md))`(`filterBitmap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md))`(`repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the number of times to repeat the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Start the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/graphics/drawable/AnimatedImageDrawable.md))`()` Stop the animation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAnimationCallback](../android/graphics/drawable/AnimatedImageDrawable.md))`(`callback:` ` [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md)`)` Removes the specified animation callback. |

| Protected methods ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](../android/graphics/drawable/AnimatedImageDrawable.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](../android/graphics/drawable/Drawable.md) |----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](../android/graphics/drawable/Drawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` Applies the specified theme to this Drawable and its children. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](../android/graphics/drawable/Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](../android/graphics/drawable/Drawable.md))`()` Removes the color filter for this drawable. <br /> | | [Rect](../android/graphics/Rect.md) | [copyBounds](../android/graphics/drawable/Drawable.md))`()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](../android/graphics/drawable/Drawable.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromPath](../android/graphics/drawable/Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable from file path name. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromResourceStream](../android/graphics/drawable/Drawable.md))`(`res:` ` [Resources](../android/content/res/Resources.md)?`, `value:` ` [TypedValue](../android/util/TypedValue.md)?`, `is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromResourceStream](../android/graphics/drawable/Drawable.md))`(`res:` ` [Resources](../android/content/res/Resources.md)?`, `value:` ` [TypedValue](../android/util/TypedValue.md)?`, `is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromStream](../android/graphics/drawable/Drawable.md))`(`is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXml](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXml](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXmlInner](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXmlInner](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | [Rect](../android/graphics/Rect.md) | [getBounds](../android/graphics/drawable/Drawable.md))`()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](../android/graphics/drawable/Drawable.md))`()` Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](../android/graphics/drawable/Drawable.md))`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](../android/graphics/drawable/Drawable.md)) or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](../android/graphics/drawable/Drawable.md))`()` Return a [ConstantState](../android/graphics/drawable/Drawable.ConstantState.md) instance that holds the shared state of this Drawable. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [getCurrent](../android/graphics/drawable/Drawable.md))`()` <br /> | | [Rect](../android/graphics/Rect.md) | [getDirtyBounds](../android/graphics/drawable/Drawable.md))`()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](../android/graphics/drawable/Drawable.md))`(`outRect:` ` [Rect](../android/graphics/Rect.md)`)` Populates `outRect` with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](../android/graphics/drawable/Drawable.md))`()` Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](../android/graphics/drawable/Drawable.md))`()` Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](../android/graphics/drawable/Drawable.md))`()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](../android/graphics/drawable/Drawable.md))`()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Insets](../android/graphics/Insets.md) | [getOpticalInsets](../android/graphics/drawable/Drawable.md))`()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](../android/graphics/drawable/Drawable.md))`(`outline:` ` [Outline](../android/graphics/Outline.md)`)` Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](../android/view/ViewOutlineProvider.md) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](../android/graphics/drawable/Drawable.md))`(`padding:` ` [Rect](../android/graphics/Rect.md)`)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](../android/graphics/drawable/Drawable.md))`()` Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android/graphics/Region.md)? | [getTransparentRegion](../android/graphics/drawable/Drawable.md))`()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](../android/graphics/drawable/Drawable.md))`()` Indicates whether this drawable has at least one state spec explicitly specifying [android.R.attr#state_focused](../android/R.attr.md). Note: A View uses a [Drawable](../android/graphics/drawable/Drawable.md) instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its [android.R.attr#state_focused](../android/R.attr.md) to make sure the user knows which view is holding the focus. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](../android/graphics/drawable/Drawable.md))`()` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](../android/graphics/drawable/Drawable.md))`()` Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android/graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](../android/graphics/drawable/Drawable.md))`()` Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/graphics/drawable/Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](../android/graphics/drawable/Drawable.md))`()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [mutate](../android/graphics/drawable/Drawable.md))`()` Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](../android/graphics/drawable/Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Override this in your subclass to change appearance if you vary based on level. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](../android/graphics/drawable/Drawable.md))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Override this in your subclass to change appearance if you recognize the specified state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](../android/graphics/drawable/Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](../android/graphics/drawable/Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](../android/graphics/drawable/Drawable.md))`(`what:` ` [Runnable](../java/lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](../android/graphics/drawable/Drawable.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](../android/graphics/drawable/Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](../android/graphics/drawable/Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](../android/graphics/drawable/Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](../android/graphics/drawable/Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) which constructs a [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](../android/graphics/drawable/Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](../android/graphics/drawable/Drawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](../android/graphics/drawable/Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](../android/graphics/drawable/Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](../android/graphics/drawable/Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](../android/graphics/drawable/Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](../android/graphics/drawable/Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](../android/graphics/drawable/Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](../android/graphics/drawable/Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](../android/graphics/drawable/Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)). To clear the tint, pass `null` to [setTintList(android.content.res.ColorStateList)](../android/graphics/drawable/Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](../android/graphics/drawable/Drawable.md))`(`blendMode:` ` [BlendMode](../android/graphics/BlendMode.md)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android/graphics/BlendMode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](../android/graphics/drawable/Drawable.md))`(`tint:` ` [ColorStateList](../android/content/res/ColorStateList.md)?`)` Specifies tint color for this drawable as a color state list. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](../android/graphics/drawable/Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)) overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](../android/graphics/drawable/Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](../android/graphics/drawable/Drawable.md))`(`what:` ` [Runnable](../java/lang/Runnable.md)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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

Pass this to [setRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md)) to repeat infinitely.

[Animatable2.AnimationCallback.onAnimationEnd](../android/graphics/drawable/Animatable2.AnimationCallback.md)) will never be called unless there is an error. 

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
| `canvas` | [Canvas](../android/graphics/Canvas.md): This value cannot be `null`. |

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
| [ColorFilter](../android/graphics/ColorFilter.md)? | This value may be `null`. |

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

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in [android.graphics.PixelFormat](../android/graphics/PixelFormat.md): [android.graphics.PixelFormat#UNKNOWN](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android/graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android/graphics/PixelFormat.md).

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method [resolveOpacity](../android/graphics/drawable/Drawable.md)) to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the [setAlpha](../android/graphics/drawable/Drawable.md)) or #setColorFilter methods. Some subclasses, such as [BitmapDrawable](../android/graphics/drawable/BitmapDrawable.md), [ColorDrawable](../android/graphics/drawable/ColorDrawable.md), and [GradientDrawable](../android/graphics/drawable/GradientDrawable.md), do account for the value of [setAlpha](../android/graphics/drawable/Drawable.md)), but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.PixelFormat#UNKNOWN](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android/graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android/graphics/PixelFormat.md) |

### getRepeatCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRepeatCount(): Int
```

Retrieve the number of times the animation will repeat.

By default, the repeat count in the encoded data is respected. If the value is [REPEAT_INFINITE](../android/graphics/drawable/AnimatedImageDrawable.md), the animation will repeat as long as it is displayed. If the value is `0`, it will play once.

Calling [setRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md)) will make future calls to this method return the value passed to [setRepeatCount](../android/graphics/drawable/AnimatedImageDrawable.md)). 

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
| `r` | [Resources](../android/content/res/Resources.md): Resources used to resolve attribute values This value cannot be `null`. |
| `parser` | [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md): XML parser from which to inflate this Drawable This value cannot be `null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md): Base set of attribute values This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: Theme to apply, may be null |

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

When this drawable is created, this will return `false`. A client needs to call [start](../android/graphics/drawable/AnimatedImageDrawable.md)) to start the animation.

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
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new resolved layout direction Value is [android.view.View#LAYOUT_DIRECTION_LTR](../android/view/View.md), or [android.view.View#LAYOUT_DIRECTION_RTL](../android/view/View.md) |

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
| `callback` | [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md): This value cannot be `null`. |

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

**Note:** Setting a non-`null` color filter disables [tint](../android/graphics/drawable/Drawable.md)).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](../android/graphics/ColorFilter.md)?: This value may be `null`. |

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

By default, the repeat count in the encoded data is respected. If set to [REPEAT_INFINITE](../android/graphics/drawable/AnimatedImageDrawable.md), the animation will repeat as long as it is displayed. If the value is `0`, the animation will play once.

This call replaces the current repeat count. If the encoded data specified a repeat count of `2` (meaning that [getRepeatCount()](../android/graphics/drawable/AnimatedImageDrawable.md)) returns `2`, the animation will play three times. Calling `setRepeatCount(1)` will result in playing only twice and [getRepeatCount()](../android/graphics/drawable/AnimatedImageDrawable.md)) returning `1`.

If the animation is already playing, the iterations that have already occurred count towards the new count. If the animation has already repeated the appropriate number of times (or more), it will finish its current iteration and then stop.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.graphics.drawable.AnimatedImageDrawable#REPEAT_INFINITE](../android/graphics/drawable/AnimatedImageDrawable.md) or greater |

### start

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Start the animation.

Does nothing if the animation is already running. If the animation is stopped, this will reset it.

When the drawable is drawn, starting the animation, [Animatable2.AnimationCallback.onAnimationStart](../android/graphics/drawable/Animatable2.AnimationCallback.md)) will be called. 

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
| `callback` | [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md): This value cannot be `null`. |

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
| `bounds` | [Rect](../android/graphics/Rect.md): This value cannot be `null`. |
