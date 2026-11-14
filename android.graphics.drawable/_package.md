# android.graphics.drawable

# android.graphics.drawable

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [Animatable](Animatable.md) | Interface that drawables supporting animations should implement. |
| --- | --- |
| [Animatable2](Animatable2.md) | Abstract class that drawables supporting animations and callbacks should extend. |
| [Callback](../android/graphics/drawable/Drawable.Callback.md) | Implement this interface if you want to create an animated drawable that extends [Drawable](Drawable.md). |
| [OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md) | Implement this interface to receive a callback when [loadDrawableAsync](Icon.md))is finished and your Drawable is ready. |
| --- | --- |

## Classes

| [AdaptiveIconDrawable](AdaptiveIconDrawable.md) | This class can also be created via XML inflation using`<adaptive-icon>`tag in addition to dynamic creation. |
| --- | --- |
| [AnimatedImageDrawable](AnimatedImageDrawable.md) | [Drawable](Drawable.md) for drawing animated images (like GIF). |
| [AnimatedStateListDrawable](AnimatedStateListDrawable.md) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. |
| [AnimatedVectorDrawable](AnimatedVectorDrawable.md) | This class animates properties of a [android.graphics.drawable.VectorDrawable](VectorDrawable.md) with animations defined using [android.animation.ObjectAnimator](../android.animation/ObjectAnimator.md) or [android.animation.AnimatorSet](../android.animation/AnimatorSet.md). |
| --- | --- |
| [AnimationDrawable](AnimationDrawable.md) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. |
| [BitmapDrawable](BitmapDrawable.md) | A Drawable that wraps a bitmap and can be tiled, stretched, or aligned. |
| [ClipDrawable](ClipDrawable.md) | A Drawable that clips another Drawable based on this Drawable's current level value. |
| --- | --- |
| [ColorDrawable](ColorDrawable.md) | A specialized Drawable that fills the Canvas with a specified color. |
| [ColorStateListDrawable](ColorStateListDrawable.md) | A Drawable that manages a [ColorDrawable](ColorDrawable.md) to make it stateful and backed by a [ColorStateList](../android.content.res/ColorStateList.md). |
| [Drawable](Drawable.md) | A Drawable is a general abstraction for "something that can be drawn. |
| --- | --- |
| [DrawableContainer](DrawableContainer.md) | A helper class that contains several [Drawable](Drawable.md) s and selects which one to use. |
| [DrawableWrapper](DrawableWrapper.md) | Drawable container with only one child element. |
| [GradientDrawable](GradientDrawable.md) | A Drawable with a color gradient for buttons, backgrounds, etc. |
| --- | --- |
| [Icon](Icon.md) | An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors). |
| [InsetDrawable](InsetDrawable.md) | A Drawable that insets another Drawable by a specified distance or fraction of the content bounds. |
| [LayerDrawable](LayerDrawable.md) | A Drawable that manages an array of other Drawables. |
| --- | --- |
| [LevelListDrawable](LevelListDrawable.md) | A resource that manages a number of alternate Drawables, each assigned a maximum numerical value. |
| [NinePatchDrawable](NinePatchDrawable.md) | A resizeable bitmap, with stretchable areas that you define. |
| [PaintDrawable](PaintDrawable.md) | Drawable that draws its bounds in the given paint, with optional rounded corners. |
| --- | --- |
| [PictureDrawable](PictureDrawable.md) | Drawable subclass that wraps a Picture, allowing the picture to be used wherever a Drawable is supported. |
| [RippleDrawable](RippleDrawable.md) | Drawable that shows a ripple effect in response to state changes. |
| [RotateDrawable](RotateDrawable.md) | A Drawable that can rotate another Drawable based on the current level value. |
| --- | --- |
| [ScaleDrawable](ScaleDrawable.md) | A Drawable that changes the size of another Drawable based on its current level value. |
| [ShapeDrawable](ShapeDrawable.md) | A Drawable object that draws primitive shapes. |
| [StateListDrawable](StateListDrawable.md) | Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value. |
| --- | --- |
| [TransitionDrawable](TransitionDrawable.md) | An extension of LayerDrawables that is intended to cross-fade between the first and second layer. |
| [VectorDrawable](VectorDrawable.md) | This lets you create a drawable based on an XML vector graphic. |
